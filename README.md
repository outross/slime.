pragma solidity ^0.8.0

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract Sugmon is ERC20, Ownable {
    uint256 public constant MAX_SUPPLY = 4000000;

    constructor() ERC20("Sugmon", "SG") {
        _mint(msg.sender, MAX_SUPPLY);
    }

    function mint(address to, uint256 amount) public onlyOwner {
        require(totalSupply() + amount <= MAX_SUPPLY, "Exceeds max total supply");
        _mint(to, amount);# slime.
beta 
